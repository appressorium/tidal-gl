# tidal-gl
Tidal, but with OpenGL
relies on glut
relies on opengl

??

https://github.com/ekmett/gl
https://github.com/ekmett/linear
https://github.com/dpwright/dpwright.github.com/blob/source/posts/2015-03-25-the-haskell-gl-package.lhs

[1 of 1] Compiling Main             ( haskell-gl.lhs, haskell-gl.o )

-- resolved at least via diff
haskell-gl.lhs:390:8:
    Couldn't match expected type ‘(Resources -> IO ())
                                  -> (IORef (M44 GLfloat) -> Int -> Int -> IO ()) -> IO ()’
                with actual type ‘IO ()’
    The function ‘loop’ is applied to three arguments,
    but its type ‘DemoState -> IO ()’ has only one
    In a stmt of a 'do' block: loop defaultState cleanup resize
    In the expression: do { loop defaultState cleanup resize }

-- unresolved
haskell-gl.lhs:409:51:
    Couldn't match type ‘V3 (V3 GLfloat)’ with ‘Maybe (t0 (t0 a0))’
    Expected type: Maybe (t0 (t0 a0))
      Actual type: Linear.Matrix.M33 GLfloat
    Relevant bindings include
      normalMat :: t0 (t0 a0) (bound at haskell-gl.lhs:409:8)
    In the third argument of ‘maybe’, namely ‘inverseMat’
    In the expression: maybe identity distribute inverseMat

